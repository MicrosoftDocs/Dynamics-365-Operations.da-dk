---
title: Konfigurere en mailbeskedprofil
description: Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555301"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="e4f03-103">Konfigurere en profil for mailbesked</span><span class="sxs-lookup"><span data-stu-id="e4f03-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4f03-104">Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4f03-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4f03-105">Når du opretter kanaler, kan du oprette en mailbeskedprofil.</span><span class="sxs-lookup"><span data-stu-id="e4f03-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="e4f03-106">På den måde kan der sendes e-mails til kunder for forskellige transaktionshændelser, som f.eks. ordreoprettelse, ordreforsendelsesstatus og betalingsfejl.</span><span class="sxs-lookup"><span data-stu-id="e4f03-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="e4f03-107">Du kan finde yderligere oplysninger om mailkonfiguration i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e4f03-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="e4f03-108">Oprette en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="e4f03-108">Create an email notification profile</span></span>

<span data-ttu-id="e4f03-109">Benyt følgende fremgangsmåde for at oprette en mailbeskedprofil.</span><span class="sxs-lookup"><span data-stu-id="e4f03-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="e4f03-110">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="e4f03-111">Klik på **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e4f03-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="e4f03-112">Angiv et navn, der identificerer profilen, i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="e4f03-113">Indtast en relevant beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="e4f03-114">Angiv parameteren **Aktiv** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="e4f03-115">Opret en mailskabelon</span><span class="sxs-lookup"><span data-stu-id="e4f03-115">Create an email template</span></span>

<span data-ttu-id="e4f03-116">Før en type mailbesked kan aktiveres, skal du oprette en mailskabelon til organisationen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e4f03-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="e4f03-117">Denne skabelon definerer mailemnet, afsenderen, standardsproget og mailbrødteksten for hvert sprog, du vil understøtte.</span><span class="sxs-lookup"><span data-stu-id="e4f03-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="e4f03-118">Benyt følgende fremgangsmåde for at oprette en mailskabelon.</span><span class="sxs-lookup"><span data-stu-id="e4f03-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="e4f03-119">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="e4f03-120">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e4f03-121">I feltet **Mail-id** sal du angive et id, der kan hjælpe med at identificere denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="e4f03-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="e4f03-122">Indtast navnet på afsenderen i feltet **Afsenders e-mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="e4f03-123">Indtast en meningsfuld beskrivelse i feltet **E-mail-beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="e4f03-124">I feltet **Afsenders e-mailadresse** skal du angive afsenderens mailadresse.</span><span class="sxs-lookup"><span data-stu-id="e4f03-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="e4f03-125">Vælg et standardsprog til mailskabelonen under **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="e4f03-126">Standardsproget bruges, når der ikke findes en lokaliseret skabelon for det angivne sprog.</span><span class="sxs-lookup"><span data-stu-id="e4f03-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="e4f03-127">Udvid sektionen **E-mailbeskedens indhold**, og vælg **Ny** for at oprette skabelonindholdet.</span><span class="sxs-lookup"><span data-stu-id="e4f03-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="e4f03-128">Vælg sproget for hvert indholdselement, og angiv emnelinjen i mailen.</span><span class="sxs-lookup"><span data-stu-id="e4f03-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="e4f03-129">Hvis der skal være indhold i mailen, skal du sørge for at markere afkrydsningsfeltet **Har indhold**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="e4f03-130">Vælg **E-mail-besked** i handlingsruden for at oprette en skabelon til mailindholdet.</span><span class="sxs-lookup"><span data-stu-id="e4f03-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="e4f03-131">Følgende billede viser eksempler på indstillinger for mailskabeloner.</span><span class="sxs-lookup"><span data-stu-id="e4f03-131">The following image shows some example email template settings.</span></span>

![Mailskabelonindstillinger](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="e4f03-133">Opret en mailhændelse</span><span class="sxs-lookup"><span data-stu-id="e4f03-133">Create an email event</span></span>

<span data-ttu-id="e4f03-134">Benyt følgende fremgangsmåde for at oprette en mailhændelse.</span><span class="sxs-lookup"><span data-stu-id="e4f03-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="e4f03-135">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="e4f03-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e4f03-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="e4f03-137">Vælg mailskabelonen fra rullelisten **Mail-id**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="e4f03-138">Vælg den relevante **E-mailbeskedtype** på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="e4f03-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="e4f03-139">Marker afkrydsningsfeltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="e4f03-140">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e4f03-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e4f03-141">Følgende billede viser eksempler på indstillinger for hændelsesbeskeder.</span><span class="sxs-lookup"><span data-stu-id="e4f03-141">The following image shows some example event notification settings.</span></span>

![Indstillinger for hændelsesbesked](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="e4f03-143">Næste trin</span><span class="sxs-lookup"><span data-stu-id="e4f03-143">Next steps</span></span>

<span data-ttu-id="e4f03-144">Før du kan sende mails, skal du konfigurere tjenesten til udgående mail og konfigurere et batchjob.</span><span class="sxs-lookup"><span data-stu-id="e4f03-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="e4f03-145">Du kan få flere oplysninger under [Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e4f03-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="e4f03-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e4f03-146">Additional resources</span></span>

[<span data-ttu-id="e4f03-147">Konfigurere og sende mail</span><span class="sxs-lookup"><span data-stu-id="e4f03-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e4f03-148">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="e4f03-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e4f03-149">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="e4f03-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="e4f03-150">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="e4f03-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
