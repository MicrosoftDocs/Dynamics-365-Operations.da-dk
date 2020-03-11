---
title: Konfigurere en callcenter-kanal
description: Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057873"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="30412-103">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="30412-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="30412-104">Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30412-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30412-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="30412-105">Overview</span></span>

<span data-ttu-id="30412-106">I Dynamics 365 Commerce er et callcenter en type kanal, som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="30412-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="30412-107">Hvis du definerer en kanal til dit callcenter, kan systemet binde specifikke data og ordrebehandlingstandarder til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="30412-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="30412-108">Et firma kan definere flere callcenter-kanaler i Commerce.</span><span class="sxs-lookup"><span data-stu-id="30412-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="30412-109">Før du opretter en ny callcenter-kanal, skal du sikre dig, at du har fuldført [forudsætningerne for kanalopsætning](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="30412-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="30412-110">Oprette og konfigurere en ny callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="30412-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="30412-111">Følg disse trin for at oprette en ny callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="30412-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="30412-112">Gå til **Moduler \> Kanaler \> Callcentre \> Alle callcentre** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="30412-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="30412-113">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="30412-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="30412-114">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="30412-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="30412-115">Vælg den relevante **juridiske enhed** fra rullelisten.</span><span class="sxs-lookup"><span data-stu-id="30412-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="30412-116">Vælg det relevante **Lagersted** fra rullelisten.</span><span class="sxs-lookup"><span data-stu-id="30412-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="30412-117">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="30412-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="30412-118">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="30412-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="30412-119">Angiv en oplysningskode for **Prisændring**.</span><span class="sxs-lookup"><span data-stu-id="30412-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="30412-120">Bemærk! Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="30412-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="30412-121">Angiv en oplysningskode for **Venteposition**.</span><span class="sxs-lookup"><span data-stu-id="30412-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="30412-122">Bemærk! Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="30412-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="30412-123">Angiv en oplysningskode for **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="30412-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="30412-124">Bemærk! Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="30412-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="30412-125">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="30412-125">Select **Save**.</span></span>

<span data-ttu-id="30412-126">Følgende billede viser oprettelsen af en ny callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="30412-126">The following image shows the creation of a new call center channel.</span></span>

![Ny callcenter-kanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="30412-128">Følgende billede viser et eksempel på en callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="30412-128">The following image shows an example call center channel.</span></span>

![Eksempel på call center-kanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="30412-130">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="30412-130">Additional channel setup</span></span>

<span data-ttu-id="30412-131">Yderligere opgaver, der kræves til konfiguration af callcenter-kanalen, omfatter opsætning af betalingsmetoder og leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="30412-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="30412-132">Følgende billede viser opsætningsindstillinger til **Leveringsmetoder** og **Betalingsmetoder** under fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="30412-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Yderligere handlinger til konfiguration af callcenter-kanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="30412-134">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="30412-134">Set up payment methods</span></span>

<span data-ttu-id="30412-135">Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="30412-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="30412-136">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="30412-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="30412-137">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="30412-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="30412-138">Vælg den ønskede betalingsmetode i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="30412-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="30412-139">Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.</span><span class="sxs-lookup"><span data-stu-id="30412-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="30412-140">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="30412-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="30412-141">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="30412-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="30412-142">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="30412-142">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="30412-144">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="30412-144">Set up modes of delivery</span></span>

<span data-ttu-id="30412-145">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="30412-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="30412-146">Udfør følgende trin for at ændre eller tilføje en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="30412-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="30412-147">Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="30412-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="30412-148">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.</span><span class="sxs-lookup"><span data-stu-id="30412-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="30412-149">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen.</span><span class="sxs-lookup"><span data-stu-id="30412-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="30412-150">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="30412-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="30412-151">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="30412-151">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="30412-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="30412-153">Additional resources</span></span>

[<span data-ttu-id="30412-154">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="30412-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="30412-155">Funktionalitet til callcenter-salg</span><span class="sxs-lookup"><span data-stu-id="30412-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="30412-156">Konfigurere indstillinger for callcenter-ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="30412-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="30412-157">Callcenter-kataloger</span><span class="sxs-lookup"><span data-stu-id="30412-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="30412-158">Konfigurere og arbejde med advarsler om svindel</span><span class="sxs-lookup"><span data-stu-id="30412-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="30412-159">Oprette kontinuitetsprogrammer for callcentre</span><span class="sxs-lookup"><span data-stu-id="30412-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
