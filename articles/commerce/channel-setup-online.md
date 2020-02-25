---
title: Konfigurere en onlinekanal
description: Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002421"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="9e120-103">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="9e120-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e120-104">Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e120-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e120-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="9e120-105">Overview</span></span>

<span data-ttu-id="9e120-106">Dynamics 365 Commerce understøtter flere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="9e120-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="9e120-107">Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="9e120-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="9e120-108">Onlinebutikker giver kunderne mulighed for at købe produkter fra detailhandlerens onlinebutik ud over fra detailhandlerens fysiske butik.</span><span class="sxs-lookup"><span data-stu-id="9e120-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="9e120-109">Hvis du vil oprette en onlinebutik i Commerce, skal du først oprette en onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="9e120-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="9e120-110">Før du opretter en ny onlinekanal, skal du sikre dig, at du har fuldført [forudsætningerne for kanalopsætning](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9e120-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="9e120-111">Oprette og konfigurere en ny onlinekanal</span><span class="sxs-lookup"><span data-stu-id="9e120-111">Create and configure a new online channel</span></span>

<span data-ttu-id="9e120-112">Følg disse trin for at oprette en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="9e120-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="9e120-113">Gå til **Moduler \>Kanaler \> Onlinebutikker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="9e120-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="9e120-114">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9e120-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e120-115">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9e120-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="9e120-116">Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="9e120-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="9e120-117">Angiv det relevante **Lagersted** på rullelisten Lagersted.</span><span class="sxs-lookup"><span data-stu-id="9e120-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="9e120-118">Vælg den relevante tidszone i feltet **Lagertidszone**.</span><span class="sxs-lookup"><span data-stu-id="9e120-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="9e120-119">Vælg den relevante valuta i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="9e120-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="9e120-120">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="9e120-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="9e120-121">Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="9e120-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="9e120-122">Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="9e120-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="9e120-123">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="9e120-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="9e120-124">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9e120-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e120-125">Følgende billede viser oprettelsen af en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="9e120-125">The following image shows the creation of a new online channel.</span></span>

![Ny onlinekanal](media/channel-setup-online-1.png)

<span data-ttu-id="9e120-127">Følgende billede viser et eksempel på en onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="9e120-127">The following image shows an example online channel.</span></span>

![Eksempel på onlinekanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="9e120-129">Konfigurer sprog</span><span class="sxs-lookup"><span data-stu-id="9e120-129">Set up languages</span></span>

<span data-ttu-id="9e120-130">Hvis dit e-handels-websted skal understøtte flere sprog, skal du udvide afsnittet **Sprog** og tilføje flere sprog efter behov.</span><span class="sxs-lookup"><span data-stu-id="9e120-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="9e120-131">Konfigurere betalingskonto</span><span class="sxs-lookup"><span data-stu-id="9e120-131">Set up payment account</span></span>

<span data-ttu-id="9e120-132">Du kan tilføje en tredjepartsbetalingsudbyder i sektionen **Betalingskonto**.</span><span class="sxs-lookup"><span data-stu-id="9e120-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="9e120-133">Du kan få oplysninger om konfiguration af en Adyen-betalingsforbindelse i [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="9e120-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="9e120-134">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="9e120-134">Additional channel set up</span></span>

<span data-ttu-id="9e120-135">Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, leveringsmetoder og gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="9e120-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="9e120-136">Følgende billede viser opsætningsindstillinger til **Leveringsmetoder**, **Betalingsmetoder** og **Gruppetildeling for opfyldelse** under fanen **Opsætning** .</span><span class="sxs-lookup"><span data-stu-id="9e120-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Yderligere handlinger til konfiguration af onlinekanal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="9e120-138">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="9e120-138">Set up payment methods</span></span>

<span data-ttu-id="9e120-139">Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="9e120-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="9e120-140">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="9e120-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="9e120-141">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9e120-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e120-142">Vælg den ønskede betalingsmetode i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="9e120-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="9e120-143">Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.</span><span class="sxs-lookup"><span data-stu-id="9e120-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="9e120-144">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="9e120-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="9e120-145">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9e120-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e120-146">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="9e120-146">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="9e120-148">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="9e120-148">Set up modes of delivery</span></span>

<span data-ttu-id="9e120-149">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="9e120-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="9e120-150">Udfør følgende trin for at ændre eller tilføje en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="9e120-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="9e120-151">Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="9e120-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="9e120-152">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.</span><span class="sxs-lookup"><span data-stu-id="9e120-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="9e120-153">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen.</span><span class="sxs-lookup"><span data-stu-id="9e120-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="9e120-154">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="9e120-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="9e120-155">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="9e120-155">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="9e120-157">Konfigurer en gruppetildeling for opfyldelse</span><span class="sxs-lookup"><span data-stu-id="9e120-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="9e120-158">Gør følgende for at konfigurere en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="9e120-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="9e120-159">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.</span><span class="sxs-lookup"><span data-stu-id="9e120-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="9e120-160">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9e120-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9e120-161">Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9e120-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="9e120-162">Indtast en beskrivelse i rullelisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9e120-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="9e120-163">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9e120-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9e120-164">Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="9e120-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Konfigurer Gruppetildeling for opfyldelse](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="9e120-166">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9e120-166">Additional resources</span></span>

[<span data-ttu-id="9e120-167">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="9e120-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9e120-168">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="9e120-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9e120-169">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="9e120-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="9e120-170">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="9e120-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="9e120-171">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="9e120-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
